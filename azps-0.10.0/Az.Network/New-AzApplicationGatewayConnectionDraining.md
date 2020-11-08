---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 813569705831dcd3d8c379b3c40078184498899e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922178"
---
# <span data-ttu-id="936bf-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="936bf-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="936bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="936bf-102">SYNOPSIS</span></span>
<span data-ttu-id="936bf-103">Skapar en ny anslutning för konfiguration av backend-HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="936bf-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="936bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="936bf-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="936bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="936bf-105">DESCRIPTION</span></span>
<span data-ttu-id="936bf-106">Cmdleten **New-AzApplicationGatewayConnectionDraining** skapar en ny anslutning för konfiguration av backend-http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="936bf-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="936bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="936bf-107">EXAMPLES</span></span>

### <span data-ttu-id="936bf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="936bf-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="936bf-109">Kommandot skapar en ny konfiguration för tömning av anslutning med aktiverat värdet true och DrainTimeoutInSec angivet till 42 sekunder och lagrar det i $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="936bf-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="936bf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="936bf-110">PARAMETERS</span></span>

### <span data-ttu-id="936bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="936bf-111">-DefaultProfile</span></span>
<span data-ttu-id="936bf-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="936bf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="936bf-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="936bf-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="936bf-114">Antalet sekunder som anslutningen är aktiv.</span><span class="sxs-lookup"><span data-stu-id="936bf-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="936bf-115">Godkända värden är mellan 1 sekund och 3600 sekunder.</span><span class="sxs-lookup"><span data-stu-id="936bf-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="936bf-116">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="936bf-116">-Enabled</span></span>
<span data-ttu-id="936bf-117">Om anslutning är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="936bf-117">Whether connection draining is enabled or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="936bf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="936bf-118">CommonParameters</span></span>
<span data-ttu-id="936bf-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="936bf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="936bf-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="936bf-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="936bf-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="936bf-121">INPUTS</span></span>

### <span data-ttu-id="936bf-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="936bf-122">None</span></span>

## <span data-ttu-id="936bf-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="936bf-123">OUTPUTS</span></span>

### <span data-ttu-id="936bf-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="936bf-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="936bf-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="936bf-125">NOTES</span></span>

## <span data-ttu-id="936bf-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="936bf-126">RELATED LINKS</span></span>

[<span data-ttu-id="936bf-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="936bf-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="936bf-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="936bf-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="936bf-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="936bf-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
