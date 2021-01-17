---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424963"
---
# <span data-ttu-id="a8f02-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="a8f02-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="a8f02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8f02-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f02-103">Skapar ett nytt ASN-PNRP</span><span class="sxs-lookup"><span data-stu-id="a8f02-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="a8f02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8f02-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8f02-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8f02-105">DESCRIPTION</span></span>
<span data-ttu-id="a8f02-106">Skapar ett nytt PeerAsn-objekt för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a8f02-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="a8f02-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8f02-107">EXAMPLES</span></span>

### <span data-ttu-id="a8f02-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a8f02-108">Example 1</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="a8f02-109">Skapar en ny PeerAsn</span><span class="sxs-lookup"><span data-stu-id="a8f02-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="a8f02-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8f02-110">PARAMETERS</span></span>

### <span data-ttu-id="a8f02-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8f02-111">-AsJob</span></span>
<span data-ttu-id="a8f02-112">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="a8f02-112">Run in the background.</span></span>

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

### <span data-ttu-id="a8f02-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="a8f02-113">-ContactDetail</span></span>
<span data-ttu-id="a8f02-114">E-postadresser som används för att kontakta dig om problem arrise vanligt vis ett nätverks åtgärds Center</span><span class="sxs-lookup"><span data-stu-id="a8f02-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f02-115">-DefaultProfile</span></span>
<span data-ttu-id="a8f02-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8f02-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8f02-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8f02-117">-Name</span></span>
<span data-ttu-id="a8f02-118">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a8f02-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a8f02-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="a8f02-119">-PeerAsn</span></span>
<span data-ttu-id="a8f02-120">Resurs-ID för peer-PNRP. Använd Get-AzPeerAsn för att hämta ID.</span><span class="sxs-lookup"><span data-stu-id="a8f02-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="a8f02-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="a8f02-121">-PeerName</span></span>
<span data-ttu-id="a8f02-122">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a8f02-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a8f02-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8f02-123">-Confirm</span></span>
<span data-ttu-id="a8f02-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8f02-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8f02-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8f02-125">-WhatIf</span></span>
<span data-ttu-id="a8f02-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8f02-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8f02-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8f02-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8f02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f02-128">CommonParameters</span></span>
<span data-ttu-id="a8f02-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8f02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f02-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8f02-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f02-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8f02-131">INPUTS</span></span>

### <span data-ttu-id="a8f02-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="a8f02-132">None</span></span>

## <span data-ttu-id="a8f02-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8f02-133">OUTPUTS</span></span>

### <span data-ttu-id="a8f02-134">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="a8f02-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="a8f02-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8f02-135">NOTES</span></span>

## <span data-ttu-id="a8f02-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8f02-136">RELATED LINKS</span></span>
