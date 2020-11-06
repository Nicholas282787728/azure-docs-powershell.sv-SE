---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkUsage.md
ms.openlocfilehash: c5bb92ad330b49ff015f21ae14fab42d6583305c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585431"
---
# <span data-ttu-id="fb2cb-101">Get-AzureRmNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="fb2cb-101">Get-AzureRmNetworkUsage</span></span>

## <span data-ttu-id="fb2cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="fb2cb-103">Visar nätverks användning för en prenumeration</span><span class="sxs-lookup"><span data-stu-id="fb2cb-103">Lists network usages for a subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb2cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb2cb-104">SYNTAX</span></span>

```
Get-AzureRmNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb2cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb2cb-105">DESCRIPTION</span></span>
<span data-ttu-id="fb2cb-106">Get-AzureRmNetworkUsage cmdlet får gränser och aktuell användning för nätverks resurser.</span><span class="sxs-lookup"><span data-stu-id="fb2cb-106">The Get-AzureRmNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="fb2cb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb2cb-107">EXAMPLES</span></span>

### <span data-ttu-id="fb2cb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fb2cb-108">Example 1</span></span>
```
PS C:\> Get-AzureRmNetworkUsage -Location westcentralus

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

<span data-ttu-id="fb2cb-109">Hämtar resursernas användnings data i westcentralus region</span><span class="sxs-lookup"><span data-stu-id="fb2cb-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="fb2cb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb2cb-110">PARAMETERS</span></span>

### <span data-ttu-id="fb2cb-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="fb2cb-111">-Location</span></span>
<span data-ttu-id="fb2cb-112">Platsen där resursanvändningen tillfrågas.</span><span class="sxs-lookup"><span data-stu-id="fb2cb-112">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="fb2cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2cb-113">-DefaultProfile</span></span>
<span data-ttu-id="fb2cb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb2cb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb2cb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb2cb-115">CommonParameters</span></span>
<span data-ttu-id="fb2cb-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb2cb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb2cb-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb2cb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb2cb-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb2cb-118">INPUTS</span></span>

### <span data-ttu-id="fb2cb-119">System. String</span><span class="sxs-lookup"><span data-stu-id="fb2cb-119">System.String</span></span>

## <span data-ttu-id="fb2cb-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb2cb-120">OUTPUTS</span></span>

### <span data-ttu-id="fb2cb-121">Microsoft. Azure. commands. Networks. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="fb2cb-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="fb2cb-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb2cb-122">NOTES</span></span>

## <span data-ttu-id="fb2cb-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb2cb-123">RELATED LINKS</span></span>

