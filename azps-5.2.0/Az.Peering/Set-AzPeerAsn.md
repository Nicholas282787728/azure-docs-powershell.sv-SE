---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398248"
---
# <span data-ttu-id="abbfd-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="abbfd-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="abbfd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abbfd-102">SYNOPSIS</span></span>
<span data-ttu-id="abbfd-103">Uppdatera kontakt information</span><span class="sxs-lookup"><span data-stu-id="abbfd-103">Update Contact Information</span></span>

## <span data-ttu-id="abbfd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abbfd-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abbfd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abbfd-105">DESCRIPTION</span></span>
<span data-ttu-id="abbfd-106">Låter dig uppdatera kontakt information för en PeerAsn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="abbfd-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="abbfd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abbfd-107">EXAMPLES</span></span>

### <span data-ttu-id="abbfd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="abbfd-108">Example 1</span></span>
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

<span data-ttu-id="abbfd-109">Lägger till en e-postadress i peer-ASN</span><span class="sxs-lookup"><span data-stu-id="abbfd-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="abbfd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abbfd-110">PARAMETERS</span></span>

### <span data-ttu-id="abbfd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abbfd-111">-AsJob</span></span>
<span data-ttu-id="abbfd-112">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="abbfd-112">Run in the background.</span></span>

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

### <span data-ttu-id="abbfd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abbfd-113">-DefaultProfile</span></span>
<span data-ttu-id="abbfd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="abbfd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abbfd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abbfd-115">-InputObject</span></span>
<span data-ttu-id="abbfd-116">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="abbfd-116">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="abbfd-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abbfd-117">-Confirm</span></span>
<span data-ttu-id="abbfd-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="abbfd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abbfd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abbfd-119">-WhatIf</span></span>
<span data-ttu-id="abbfd-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="abbfd-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abbfd-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="abbfd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abbfd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abbfd-122">CommonParameters</span></span>
<span data-ttu-id="abbfd-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abbfd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abbfd-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abbfd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abbfd-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abbfd-125">INPUTS</span></span>

### <span data-ttu-id="abbfd-126">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="abbfd-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="abbfd-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abbfd-127">OUTPUTS</span></span>

### <span data-ttu-id="abbfd-128">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="abbfd-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="abbfd-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abbfd-129">NOTES</span></span>

## <span data-ttu-id="abbfd-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abbfd-130">RELATED LINKS</span></span>
