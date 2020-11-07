---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: 82a112363a561e7566b0d748d00acc75dc026ebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919580"
---
# <span data-ttu-id="78c8c-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="78c8c-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="78c8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="78c8c-103">Ta bort ASN i peer</span><span class="sxs-lookup"><span data-stu-id="78c8c-103">Remove Peer Asn</span></span>

## <span data-ttu-id="78c8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78c8c-104">SYNTAX</span></span>

### <span data-ttu-id="78c8c-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="78c8c-105">Default (Default)</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78c8c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="78c8c-106">ByName</span></span>
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78c8c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78c8c-107">DESCRIPTION</span></span>
<span data-ttu-id="78c8c-108">Ta bort en PeerAsn från abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="78c8c-108">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="78c8c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78c8c-109">EXAMPLES</span></span>

### <span data-ttu-id="78c8c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="78c8c-110">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="78c8c-111">Tar bort ASN för peer</span><span class="sxs-lookup"><span data-stu-id="78c8c-111">Removes the Peer Asn</span></span>

## <span data-ttu-id="78c8c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78c8c-112">PARAMETERS</span></span>

### <span data-ttu-id="78c8c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78c8c-113">-AsJob</span></span>
<span data-ttu-id="78c8c-114">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="78c8c-114">Run in the background.</span></span>

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

### <span data-ttu-id="78c8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c8c-115">-DefaultProfile</span></span>
<span data-ttu-id="78c8c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78c8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78c8c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="78c8c-117">-Force</span></span>
<span data-ttu-id="78c8c-118">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="78c8c-118">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="78c8c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78c8c-119">-InputObject</span></span>
<span data-ttu-id="78c8c-120">PeerAsn-objektet.</span><span class="sxs-lookup"><span data-stu-id="78c8c-120">The PeerAsn object.</span></span>

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

### <span data-ttu-id="78c8c-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="78c8c-121">-Name</span></span>
<span data-ttu-id="78c8c-122">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="78c8c-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="78c8c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78c8c-123">-PassThru</span></span>
<span data-ttu-id="78c8c-124">Returnera True om den är klar</span><span class="sxs-lookup"><span data-stu-id="78c8c-124">Return true if complete</span></span>

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

### <span data-ttu-id="78c8c-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78c8c-125">-Confirm</span></span>
<span data-ttu-id="78c8c-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78c8c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78c8c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78c8c-127">-WhatIf</span></span>
<span data-ttu-id="78c8c-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78c8c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78c8c-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78c8c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78c8c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c8c-130">CommonParameters</span></span>
<span data-ttu-id="78c8c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78c8c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c8c-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78c8c-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c8c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78c8c-133">INPUTS</span></span>

### <span data-ttu-id="78c8c-134">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="78c8c-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="78c8c-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78c8c-135">OUTPUTS</span></span>

### <span data-ttu-id="78c8c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78c8c-136">System.Boolean</span></span>

## <span data-ttu-id="78c8c-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78c8c-137">NOTES</span></span>

## <span data-ttu-id="78c8c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78c8c-138">RELATED LINKS</span></span>
