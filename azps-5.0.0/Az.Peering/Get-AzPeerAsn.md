---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325098"
---
# <span data-ttu-id="392ed-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="392ed-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="392ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="392ed-102">SYNOPSIS</span></span>
<span data-ttu-id="392ed-103">Hämtar PeerAsn-objekt från ARM.</span><span class="sxs-lookup"><span data-stu-id="392ed-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="392ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="392ed-104">SYNTAX</span></span>

### <span data-ttu-id="392ed-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="392ed-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="392ed-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="392ed-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="392ed-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="392ed-107">DESCRIPTION</span></span>
<span data-ttu-id="392ed-108">Hämtar PeerAsn för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="392ed-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="392ed-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="392ed-109">EXAMPLES</span></span>

### <span data-ttu-id="392ed-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="392ed-110">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -Name Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="392ed-111">Hämtar PeerAsn</span><span class="sxs-lookup"><span data-stu-id="392ed-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="392ed-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="392ed-112">PARAMETERS</span></span>

### <span data-ttu-id="392ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="392ed-113">-DefaultProfile</span></span>
<span data-ttu-id="392ed-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="392ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="392ed-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="392ed-115">-Name</span></span>
<span data-ttu-id="392ed-116">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="392ed-116">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="392ed-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="392ed-117">-ResourceId</span></span>
<span data-ttu-id="392ed-118">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="392ed-118">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="392ed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="392ed-119">CommonParameters</span></span>
<span data-ttu-id="392ed-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="392ed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="392ed-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="392ed-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="392ed-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="392ed-122">INPUTS</span></span>

### <span data-ttu-id="392ed-123">System. String</span><span class="sxs-lookup"><span data-stu-id="392ed-123">System.String</span></span>

## <span data-ttu-id="392ed-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="392ed-124">OUTPUTS</span></span>

### <span data-ttu-id="392ed-125">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="392ed-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="392ed-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="392ed-126">NOTES</span></span>

## <span data-ttu-id="392ed-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="392ed-127">RELATED LINKS</span></span>
