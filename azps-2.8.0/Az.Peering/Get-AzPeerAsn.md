---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e2588e1516b8b0ee41e260b27ea40ed72a199613
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919600"
---
# <span data-ttu-id="9ee2d-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="9ee2d-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="9ee2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ee2d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee2d-103">Hämtar PeerAsn-objekt från ARM.</span><span class="sxs-lookup"><span data-stu-id="9ee2d-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="9ee2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ee2d-104">SYNTAX</span></span>

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ee2d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ee2d-105">DESCRIPTION</span></span>
<span data-ttu-id="9ee2d-106">Hämtar PeerAsn för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9ee2d-106">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="9ee2d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ee2d-107">EXAMPLES</span></span>

### <span data-ttu-id="9ee2d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9ee2d-108">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -PeerName Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="9ee2d-109">Hämtar PeerAsn</span><span class="sxs-lookup"><span data-stu-id="9ee2d-109">Gets the PeerAsn</span></span>

## <span data-ttu-id="9ee2d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ee2d-110">PARAMETERS</span></span>

### <span data-ttu-id="9ee2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee2d-111">-DefaultProfile</span></span>
<span data-ttu-id="9ee2d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ee2d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ee2d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ee2d-113">-Name</span></span>
<span data-ttu-id="9ee2d-114">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="9ee2d-114">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee2d-115">CommonParameters</span></span>
<span data-ttu-id="9ee2d-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ee2d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee2d-117">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ee2d-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee2d-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ee2d-118">INPUTS</span></span>

### <span data-ttu-id="9ee2d-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="9ee2d-119">None</span></span>

## <span data-ttu-id="9ee2d-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ee2d-120">OUTPUTS</span></span>

### <span data-ttu-id="9ee2d-121">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="9ee2d-121">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="9ee2d-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ee2d-122">NOTES</span></span>

## <span data-ttu-id="9ee2d-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ee2d-123">RELATED LINKS</span></span>
