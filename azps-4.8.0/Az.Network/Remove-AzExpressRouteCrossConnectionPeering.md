---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 4309550557480211560e108489b14850672ee1f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261819"
---
# <span data-ttu-id="d5bb0-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d5bb0-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="d5bb0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="d5bb0-103">Tar bort en ExpressRoute-konfiguration för flera kors anslutningar.</span><span class="sxs-lookup"><span data-stu-id="d5bb0-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="d5bb0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5bb0-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5bb0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="d5bb0-106">Cmdleten **Remove-AzExpressRouteCrossConnectionPeering** tar bort en ExpressRoute-peering-konfiguration för flera anslutningar.</span><span class="sxs-lookup"><span data-stu-id="d5bb0-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="d5bb0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5bb0-107">EXAMPLES</span></span>

### <span data-ttu-id="d5bb0-108">Exempel 1: ta bort en peering-konfiguration från en ExpressRoute-kors anslutning</span><span class="sxs-lookup"><span data-stu-id="d5bb0-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="d5bb0-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5bb0-109">PARAMETERS</span></span>

### <span data-ttu-id="d5bb0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5bb0-110">-DefaultProfile</span></span>
<span data-ttu-id="d5bb0-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5bb0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5bb0-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d5bb0-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="d5bb0-113">ExpressRoute-kors anslutningen som innehåller peering-konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d5bb0-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5bb0-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d5bb0-114">-Force</span></span>
<span data-ttu-id="d5bb0-115">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="d5bb0-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d5bb0-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="d5bb0-116">-Name</span></span>
<span data-ttu-id="d5bb0-117">Namnet på peering-konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d5bb0-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="d5bb0-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="d5bb0-118">-PeerAddressType</span></span>
<span data-ttu-id="d5bb0-119">Peering-adress familjen</span><span class="sxs-lookup"><span data-stu-id="d5bb0-119">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5bb0-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d5bb0-120">-Confirm</span></span>
<span data-ttu-id="d5bb0-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d5bb0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5bb0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5bb0-122">-WhatIf</span></span>
<span data-ttu-id="d5bb0-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d5bb0-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5bb0-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d5bb0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5bb0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5bb0-125">CommonParameters</span></span>
<span data-ttu-id="d5bb0-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5bb0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5bb0-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5bb0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5bb0-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5bb0-128">INPUTS</span></span>

### <span data-ttu-id="d5bb0-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d5bb0-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="d5bb0-130">Parametern ' ExpressRouteCrossConnection ' godkänner värdet av typen ' PSExpressRouteCrossConnection ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d5bb0-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="d5bb0-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5bb0-131">OUTPUTS</span></span>

### <span data-ttu-id="d5bb0-132">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d5bb0-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="d5bb0-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5bb0-133">NOTES</span></span>

## <span data-ttu-id="d5bb0-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5bb0-134">RELATED LINKS</span></span>

[<span data-ttu-id="d5bb0-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d5bb0-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="d5bb0-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d5bb0-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](./Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="d5bb0-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d5bb0-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="d5bb0-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d5bb0-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
