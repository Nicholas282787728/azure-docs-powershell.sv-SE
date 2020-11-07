---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: 5ce29456e79755758989f208802e2850642fdcd7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919584"
---
# <span data-ttu-id="1807d-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="1807d-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="1807d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1807d-102">SYNOPSIS</span></span>
<span data-ttu-id="1807d-103">Skapar ett nytt ASN-PNRP</span><span class="sxs-lookup"><span data-stu-id="1807d-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="1807d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1807d-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -Email <String[]> -Phone <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1807d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1807d-105">DESCRIPTION</span></span>
<span data-ttu-id="1807d-106">Skapar ett nytt PeerAsn-objekt för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1807d-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="1807d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1807d-107">EXAMPLES</span></span>

### <span data-ttu-id="1807d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1807d-108">Example 1</span></span>
```powershell
PS C:> New-AzPeerAsn -Name Contoso65050 -PeerName Contoso -PeerAsn 65050 -Emails noc@contoso.com -Phone "888-888-8889"

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="1807d-109">Skapar en ny PeerAsn</span><span class="sxs-lookup"><span data-stu-id="1807d-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="1807d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1807d-110">PARAMETERS</span></span>

### <span data-ttu-id="1807d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1807d-111">-AsJob</span></span>
<span data-ttu-id="1807d-112">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="1807d-112">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1807d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1807d-113">-DefaultProfile</span></span>
<span data-ttu-id="1807d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1807d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1807d-115">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="1807d-115">-Email</span></span>
<span data-ttu-id="1807d-116">E-</span><span class="sxs-lookup"><span data-stu-id="1807d-116">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1807d-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="1807d-117">-Name</span></span>
<span data-ttu-id="1807d-118">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="1807d-118">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1807d-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="1807d-119">-PeerAsn</span></span>
<span data-ttu-id="1807d-120">Resurs-ID för peer-PNRP. Använd Get-AzPeerAsn för att hämta ID.</span><span class="sxs-lookup"><span data-stu-id="1807d-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1807d-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="1807d-121">-PeerName</span></span>
<span data-ttu-id="1807d-122">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="1807d-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1807d-123">-Telefon</span><span class="sxs-lookup"><span data-stu-id="1807d-123">-Phone</span></span>
<span data-ttu-id="1807d-124">Telefonnr</span><span class="sxs-lookup"><span data-stu-id="1807d-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1807d-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1807d-125">-Confirm</span></span>
<span data-ttu-id="1807d-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1807d-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1807d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1807d-127">-WhatIf</span></span>
<span data-ttu-id="1807d-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1807d-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1807d-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1807d-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1807d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1807d-130">CommonParameters</span></span>
<span data-ttu-id="1807d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1807d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1807d-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1807d-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1807d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1807d-133">INPUTS</span></span>

### <span data-ttu-id="1807d-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="1807d-134">None</span></span>

## <span data-ttu-id="1807d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1807d-135">OUTPUTS</span></span>

### <span data-ttu-id="1807d-136">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="1807d-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="1807d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1807d-137">NOTES</span></span>

## <span data-ttu-id="1807d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1807d-138">RELATED LINKS</span></span>
