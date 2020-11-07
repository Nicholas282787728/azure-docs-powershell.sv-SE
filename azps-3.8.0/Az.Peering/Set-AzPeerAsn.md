---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: 7931b993ff8374a84b0c2e963b8d615ce7a252fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927710"
---
# <span data-ttu-id="7ce13-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="7ce13-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="7ce13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ce13-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce13-103">Uppdatera kontakt information</span><span class="sxs-lookup"><span data-stu-id="7ce13-103">Update Contact Information</span></span>

## <span data-ttu-id="7ce13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ce13-104">SYNTAX</span></span>

### <span data-ttu-id="7ce13-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="7ce13-105">ByName (Default)</span></span>
```
Set-AzPeerAsn [-Name] <String> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ce13-106">Vis</span><span class="sxs-lookup"><span data-stu-id="7ce13-106">Default</span></span>
```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ce13-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ce13-107">DESCRIPTION</span></span>
<span data-ttu-id="7ce13-108">Låter dig uppdatera kontakt information för en PeerAsn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7ce13-108">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="7ce13-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ce13-109">EXAMPLES</span></span>

### <span data-ttu-id="7ce13-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7ce13-110">Example 1</span></span>
```powershell
#Get the Peer ASN object
PS C:> Get-AzPeerAsn -PeerName Contoso | Set-AzPeerAsn -Email noc1@contoso.com

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="7ce13-111">Lägger till en e-postadress i peer-ASN</span><span class="sxs-lookup"><span data-stu-id="7ce13-111">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="7ce13-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ce13-112">PARAMETERS</span></span>

### <span data-ttu-id="7ce13-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ce13-113">-AsJob</span></span>
<span data-ttu-id="7ce13-114">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="7ce13-114">Run in the background.</span></span>

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

### <span data-ttu-id="7ce13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce13-115">-DefaultProfile</span></span>
<span data-ttu-id="7ce13-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ce13-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ce13-117">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="7ce13-117">-Email</span></span>
<span data-ttu-id="7ce13-118">E-</span><span class="sxs-lookup"><span data-stu-id="7ce13-118">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce13-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ce13-119">-InputObject</span></span>
<span data-ttu-id="7ce13-120">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="7ce13-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ce13-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ce13-121">-Name</span></span>
<span data-ttu-id="7ce13-122">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7ce13-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce13-123">-Telefon</span><span class="sxs-lookup"><span data-stu-id="7ce13-123">-Phone</span></span>
<span data-ttu-id="7ce13-124">Telefonnr</span><span class="sxs-lookup"><span data-stu-id="7ce13-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce13-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ce13-125">-Confirm</span></span>
<span data-ttu-id="7ce13-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ce13-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ce13-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ce13-127">-WhatIf</span></span>
<span data-ttu-id="7ce13-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ce13-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ce13-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ce13-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ce13-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce13-130">CommonParameters</span></span>
<span data-ttu-id="7ce13-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ce13-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce13-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ce13-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce13-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ce13-133">INPUTS</span></span>

### <span data-ttu-id="7ce13-134">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="7ce13-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="7ce13-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ce13-135">OUTPUTS</span></span>

### <span data-ttu-id="7ce13-136">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="7ce13-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="7ce13-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ce13-137">NOTES</span></span>

## <span data-ttu-id="7ce13-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ce13-138">RELATED LINKS</span></span>
