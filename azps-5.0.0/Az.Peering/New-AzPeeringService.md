---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269267"
---
# <span data-ttu-id="637cc-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="637cc-101">New-AzPeeringService</span></span>

## <span data-ttu-id="637cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="637cc-102">SYNOPSIS</span></span>
<span data-ttu-id="637cc-103">Skapar en ny peering-tjänst.</span><span class="sxs-lookup"><span data-stu-id="637cc-103">Creates a new peering service.</span></span>

## <span data-ttu-id="637cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="637cc-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="637cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="637cc-105">DESCRIPTION</span></span>
<span data-ttu-id="637cc-106">Skapar peering service.</span><span class="sxs-lookup"><span data-stu-id="637cc-106">Creates peering service.</span></span>

## <span data-ttu-id="637cc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="637cc-107">EXAMPLES</span></span>

### <span data-ttu-id="637cc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="637cc-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="637cc-109">Skapar ett peering service-objekt med leverantör och peering-plats.</span><span class="sxs-lookup"><span data-stu-id="637cc-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="637cc-110">Använda i conjuction med `Get-AzPeeringServiceProvider` och `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="637cc-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="637cc-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="637cc-111">PARAMETERS</span></span>

### <span data-ttu-id="637cc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="637cc-112">-AsJob</span></span>
<span data-ttu-id="637cc-113">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="637cc-113">Run in the background.</span></span>

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

### <span data-ttu-id="637cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="637cc-114">-DefaultProfile</span></span>
<span data-ttu-id="637cc-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="637cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="637cc-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="637cc-116">-Name</span></span>
<span data-ttu-id="637cc-117">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="637cc-117">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="637cc-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="637cc-118">-PeeringLocation</span></span>
<span data-ttu-id="637cc-119">Den fysiska platsen skiljer sig från Azure-regionen.</span><span class="sxs-lookup"><span data-stu-id="637cc-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="637cc-120">Använd Get-AzPeeringServiceLocation [-Country <country> ]</span><span class="sxs-lookup"><span data-stu-id="637cc-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="637cc-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="637cc-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="637cc-122">Peering service leverantörens namn.</span><span class="sxs-lookup"><span data-stu-id="637cc-122">The peering service provider name.</span></span>
<span data-ttu-id="637cc-123">Använda Get-AzPeeringServiceProvider cmdlet för en lista</span><span class="sxs-lookup"><span data-stu-id="637cc-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="637cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="637cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="637cc-125">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="637cc-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="637cc-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="637cc-126">-Tag</span></span>
<span data-ttu-id="637cc-127">Taggarna som ska kopplas till Microsoft InputObject-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="637cc-127">The tags to associate with the Microsoft InputObject Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="637cc-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="637cc-128">-Confirm</span></span>
<span data-ttu-id="637cc-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="637cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="637cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="637cc-130">-WhatIf</span></span>
<span data-ttu-id="637cc-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="637cc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="637cc-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="637cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="637cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="637cc-133">CommonParameters</span></span>
<span data-ttu-id="637cc-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="637cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="637cc-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="637cc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="637cc-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="637cc-136">INPUTS</span></span>

### <span data-ttu-id="637cc-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="637cc-137">None</span></span>

## <span data-ttu-id="637cc-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="637cc-138">OUTPUTS</span></span>

### <span data-ttu-id="637cc-139">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="637cc-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="637cc-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="637cc-140">NOTES</span></span>

## <span data-ttu-id="637cc-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="637cc-141">RELATED LINKS</span></span>