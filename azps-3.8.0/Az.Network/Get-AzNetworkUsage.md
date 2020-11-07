---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: e02527c0f206607ae778d6447e65a1c93c620b02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926522"
---
# <span data-ttu-id="45439-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="45439-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="45439-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45439-102">SYNOPSIS</span></span>
<span data-ttu-id="45439-103">Visar nätverks användning för en prenumeration</span><span class="sxs-lookup"><span data-stu-id="45439-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="45439-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45439-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45439-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45439-105">DESCRIPTION</span></span>
<span data-ttu-id="45439-106">Get-AzNetworkUsage cmdlet får gränser och aktuell användning för nätverks resurser.</span><span class="sxs-lookup"><span data-stu-id="45439-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="45439-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45439-107">EXAMPLES</span></span>

### <span data-ttu-id="45439-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="45439-108">Example 1</span></span>
```
PS C:\> Get-AzNetworkUsage -Location westcentralus

ResourceType : Virtual Networks
CurrentValue : 6
Limit        : 50

ResourceType : Static Public IP Addresses
CurrentValue : 1
Limit        : 20

ResourceType : Network Security Groups
CurrentValue : 2
Limit        : 100

ResourceType : Public IP Addresses
CurrentValue : 6
Limit        : 60

ResourceType : Network Interfaces
CurrentValue : 1
Limit        : 300

ResourceType : Load Balancers
CurrentValue : 1
Limit        : 100

ResourceType : Application Gateways
CurrentValue : 1
Limit        : 50

ResourceType : Route Tables
CurrentValue : 0
Limit        : 100

ResourceType : Route Filters
CurrentValue : 0
Limit        : 1000

ResourceType : Network Watchers
CurrentValue : 1
Limit        : 1

ResourceType : Packet Captures
CurrentValue : 0
Limit        : 10
```

<span data-ttu-id="45439-109">Hämtar resursernas användnings data i westcentralus region</span><span class="sxs-lookup"><span data-stu-id="45439-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="45439-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45439-110">PARAMETERS</span></span>

### <span data-ttu-id="45439-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45439-111">-DefaultProfile</span></span>
<span data-ttu-id="45439-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45439-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45439-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="45439-113">-Location</span></span>
<span data-ttu-id="45439-114">Platsen där resursanvändningen tillfrågas.</span><span class="sxs-lookup"><span data-stu-id="45439-114">The location where resource usage is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45439-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45439-115">CommonParameters</span></span>
<span data-ttu-id="45439-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45439-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45439-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45439-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45439-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45439-118">INPUTS</span></span>

### <span data-ttu-id="45439-119">System. String</span><span class="sxs-lookup"><span data-stu-id="45439-119">System.String</span></span>

## <span data-ttu-id="45439-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45439-120">OUTPUTS</span></span>

### <span data-ttu-id="45439-121">Microsoft. Azure. commands. Networks. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="45439-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="45439-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45439-122">NOTES</span></span>

## <span data-ttu-id="45439-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45439-123">RELATED LINKS</span></span>
