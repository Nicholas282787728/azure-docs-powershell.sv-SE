---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424851"
---
# <span data-ttu-id="f25e2-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="f25e2-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="f25e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f25e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f25e2-103">Uppdatera kontakt information</span><span class="sxs-lookup"><span data-stu-id="f25e2-103">Update Contact Information</span></span>

## <span data-ttu-id="f25e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f25e2-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f25e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f25e2-105">DESCRIPTION</span></span>
<span data-ttu-id="f25e2-106">Låter dig uppdatera kontakt information för en PeerAsn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f25e2-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="f25e2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f25e2-107">EXAMPLES</span></span>

### <span data-ttu-id="f25e2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f25e2-108">Example 1</span></span>
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

<span data-ttu-id="f25e2-109">Lägger till en e-postadress i peer-ASN</span><span class="sxs-lookup"><span data-stu-id="f25e2-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="f25e2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f25e2-110">PARAMETERS</span></span>

### <span data-ttu-id="f25e2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f25e2-111">-AsJob</span></span>
<span data-ttu-id="f25e2-112">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="f25e2-112">Run in the background.</span></span>

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

### <span data-ttu-id="f25e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f25e2-113">-DefaultProfile</span></span>
<span data-ttu-id="f25e2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f25e2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f25e2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f25e2-115">-InputObject</span></span>
<span data-ttu-id="f25e2-116">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="f25e2-116">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f25e2-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f25e2-117">-Confirm</span></span>
<span data-ttu-id="f25e2-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f25e2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f25e2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f25e2-119">-WhatIf</span></span>
<span data-ttu-id="f25e2-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f25e2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f25e2-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f25e2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f25e2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f25e2-122">CommonParameters</span></span>
<span data-ttu-id="f25e2-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f25e2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f25e2-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f25e2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f25e2-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f25e2-125">INPUTS</span></span>

### <span data-ttu-id="f25e2-126">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="f25e2-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="f25e2-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f25e2-127">OUTPUTS</span></span>

### <span data-ttu-id="f25e2-128">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="f25e2-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="f25e2-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f25e2-129">NOTES</span></span>

## <span data-ttu-id="f25e2-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f25e2-130">RELATED LINKS</span></span>
