---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424896"
---
# <span data-ttu-id="5e575-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="5e575-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="5e575-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e575-102">SYNOPSIS</span></span>
<span data-ttu-id="5e575-103">Ta bort ASN i peer</span><span class="sxs-lookup"><span data-stu-id="5e575-103">Remove Peer Asn</span></span>

## <span data-ttu-id="5e575-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e575-104">SYNTAX</span></span>

### <span data-ttu-id="5e575-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="5e575-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e575-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5e575-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e575-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e575-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e575-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e575-108">DESCRIPTION</span></span>
<span data-ttu-id="5e575-109">Ta bort en PeerAsn från abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="5e575-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="5e575-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e575-110">EXAMPLES</span></span>

### <span data-ttu-id="5e575-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5e575-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="5e575-112">Tar bort ASN för peer</span><span class="sxs-lookup"><span data-stu-id="5e575-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="5e575-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e575-113">PARAMETERS</span></span>

### <span data-ttu-id="5e575-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e575-114">-AsJob</span></span>
<span data-ttu-id="5e575-115">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="5e575-115">Run in the background.</span></span>

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

### <span data-ttu-id="5e575-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e575-116">-DefaultProfile</span></span>
<span data-ttu-id="5e575-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e575-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e575-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5e575-118">-Force</span></span>
<span data-ttu-id="5e575-119">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="5e575-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="5e575-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e575-120">-InputObject</span></span>
<span data-ttu-id="5e575-121">PeerAsn-objektet.</span><span class="sxs-lookup"><span data-stu-id="5e575-121">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e575-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e575-122">-Name</span></span>
<span data-ttu-id="5e575-123">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="5e575-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e575-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e575-124">-PassThru</span></span>
<span data-ttu-id="5e575-125">Returnera True om den är klar</span><span class="sxs-lookup"><span data-stu-id="5e575-125">Return true if complete</span></span>

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

### <span data-ttu-id="5e575-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e575-126">-ResourceId</span></span>
<span data-ttu-id="5e575-127">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5e575-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e575-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e575-128">-Confirm</span></span>
<span data-ttu-id="5e575-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e575-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e575-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e575-130">-WhatIf</span></span>
<span data-ttu-id="5e575-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e575-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e575-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e575-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e575-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e575-133">CommonParameters</span></span>
<span data-ttu-id="5e575-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e575-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e575-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e575-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e575-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e575-136">INPUTS</span></span>

### <span data-ttu-id="5e575-137">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="5e575-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="5e575-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5e575-138">System.String</span></span>

## <span data-ttu-id="5e575-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e575-139">OUTPUTS</span></span>

### <span data-ttu-id="5e575-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e575-140">System.Boolean</span></span>

## <span data-ttu-id="5e575-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e575-141">NOTES</span></span>

## <span data-ttu-id="5e575-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e575-142">RELATED LINKS</span></span>
